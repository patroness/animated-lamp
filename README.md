public class For_ICT {
    public static class Time {
        private int mHour;
        private int mMinute;
        private int mSecond;
        private long mTime;

        public Time() {
            mTime = System.currentTimeMillis();
        }

        public Time(long time) {
            mTime = time;
        }
        public Time(int hour, int minute, int second) {
            mHour = hour;
            mMinute = minute;
            mSecond = second;
        }

        public void setTime(long elapsedTime) {
            mTime = elapsedTime;
        }


        public int getHour() { return (int time * 60 * 60) % 24;}

        }

        public int getMinute() {
            return (int)(mTime / (1000 * 60)) % 60;
        }

        public int getSecond() {
            return (int)(mTime / 1000) % 60;
        }

    }
    public static void main(String[] args) {
        Time time = new Time();
        System.out.printf("%dam:%d:%d\n", time.getHour(), time.getMinute(), time.getSecond());
        time.setTime(555550000);
        System.out.printf("%d:%d:%d", time.getHour(), time.getMinute(), time.getSecond());
    }
}
